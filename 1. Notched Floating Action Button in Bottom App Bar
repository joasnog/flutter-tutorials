import 'package:flutter/material.dart';

class HomePage extends StatefulWidget {
  const HomePage({super.key});

  @override
  State<HomePage> createState() => _HomePageState();
}

class _HomePageState extends State<HomePage> {
  int _index = 0;

  final List<Widget> _pages = [
    const Center(
      child: Text('Home'),
    ),
    const Center(
      child: Text('Search'),
    ),
    const Center(
      child: Text('Favorites'),
    ),
    const Center(
      child: Text('Profile'),
    ),
  ];

  void _changePage(int index) {
    setState(() {
      _index = index;
    });
  }

  BottomAppBar buildBottomAppBar() {
    return BottomAppBar(
      color: const Color(0xff00131a),
      shape: const CircularNotchedRectangle(),
      notchMargin: 8,
      child: Row(
        mainAxisAlignment: MainAxisAlignment.spaceAround,
        children: [
          IconButton(
            onPressed: () => _changePage(0),
            icon: const Icon(
              Icons.home_rounded,
              color: Colors.white,
            ),
          ),
          Padding(
            padding: const EdgeInsets.only(right: 8.0),
            child: IconButton(
              onPressed: () => _changePage(1),
              icon: const Icon(
                Icons.search_rounded,
                color: Colors.white,
              ),
            ),
          ),
          Padding(
            padding: const EdgeInsets.only(left: 8.0),
            child: IconButton(
              onPressed: () => _changePage(2),
              icon: const Icon(
                Icons.favorite_rounded,
                color: Colors.white,
              ),
            ),
          ),
          IconButton(
            onPressed: () => _changePage(3),
            icon: const Icon(
              Icons.person_rounded,
              color: Colors.white,
            ),
          ),
        ],
      ),
    );
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.grey.shade300,
      appBar: AppBar(
        title: const Text('Notched Floating Action Button'),
        backgroundColor: const Color(0xff00131a),
      ),
      body: _pages[_index],
      floatingActionButton: FloatingActionButton(
        onPressed: () {},
        backgroundColor: const Color(0xff00131a),
        child: const Icon(
          Icons.add_rounded,
        ),
      ),
      floatingActionButtonLocation: FloatingActionButtonLocation.centerDocked,
      bottomNavigationBar: buildBottomAppBar(),
    );
  }
}
