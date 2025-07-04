class User {
    String name;
    User(String name) {
        this.name = name;
    }
}

class Message {
    User sender;
    String content;

    Message(User sender, String content) {
        this.sender = sender;
        this.content = content;
    }
}

class ChatRoom {
    String roomName;
    List<Message> messages = new ArrayList<>();
    List<User> users = new ArrayList<>();

    ChatRoom(String roomName) {
        this.roomName = roomName;
    }

    void sendMessage(User user, String content) {
        Message message = new Message(user, content);
        messages.add(message);
        System.out.println(user.name + ": " + content);
    }
}
